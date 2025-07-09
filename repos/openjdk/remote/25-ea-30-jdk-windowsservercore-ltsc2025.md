## `openjdk:25-ea-30-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:cef9c38f67107891f3991184b717e55b697ba38422f644fe9817e3e4eeb0ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `openjdk:25-ea-30-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull openjdk@sha256:b0422e038fd7b9adce6d51576d28963cc7c4230c8e155c1bc238450551ce3b78
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3710846716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76703f0d4b9639b86dd0e682b66d4934a46d2f35122643c65a761bc49261265`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:09:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:28 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Jul 2025 18:09:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:37 GMT
ENV JAVA_VERSION=25-ea+30
# Wed, 09 Jul 2025 18:09:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_windows-x64_bin.zip
# Wed, 09 Jul 2025 18:09:40 GMT
ENV JAVA_SHA256=917fc8ab9ae5f7aa7aa1d45bd5a8612a2fd33d6835b9a42728532d0a14f8b42e
# Wed, 09 Jul 2025 18:09:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:10:00 GMT
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
	-	`sha256:b10375c65bf1af76d75eabda8b6510d8af93d71a5ba7a454172fdc505cfd70fa`  
		Last Modified: Wed, 09 Jul 2025 19:09:29 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5349faecc1cbbe49bfb4e55d604b75f8b9f163a9bae459e9c353e9ea0aca4ef6`  
		Last Modified: Wed, 09 Jul 2025 19:09:29 GMT  
		Size: 376.8 KB (376783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27643d5abe7ad97eef0cd4c0950b535234741f30846394208b7c20df4c9f5e11`  
		Last Modified: Wed, 09 Jul 2025 19:09:30 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9214fbf3dac7188859a0807150ef16cb5f4bf93acdf037a6d73953121f1fbe`  
		Last Modified: Wed, 09 Jul 2025 19:09:31 GMT  
		Size: 358.7 KB (358695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c673eb7d80c67dee2faacec183c6548b29b1af7b0d381ce399ff44255982f4b`  
		Last Modified: Wed, 09 Jul 2025 19:09:32 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e138e38d6089de8846ce471cdf86a0e73f73b15822bb704d2c924f90002765`  
		Last Modified: Wed, 09 Jul 2025 19:09:32 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f89f69cebf4039b93c1044ac70ec7fb3006b2fd6289f65f37351353f604b84`  
		Last Modified: Wed, 09 Jul 2025 19:09:33 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec690878083080cc7acac3b65cdcd713465d1c4f7eaf556f4fe073436b9b6c4`  
		Last Modified: Wed, 09 Jul 2025 19:10:06 GMT  
		Size: 218.9 MB (218929884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dbcf73c2e3100c89251537335af0adfe0606dc652268dc74b645e157d8eabf`  
		Last Modified: Wed, 09 Jul 2025 19:09:45 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
