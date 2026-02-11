## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:4e5b02d1fffd29cc22dda8afaddce133263964395a14669e9edcd7c9099e3e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull caddy@sha256:0b1fab1ad0f84827a4b6a1253b4dd2d39c0c6cb3a16c85486c79cb5331e44cd2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1979221351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c81865a14f9d3030678b6b0b3a674a4a9b49892d581e023603feed3b6d7dba`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:51:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:03:44 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Feb 2026 23:03:45 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Feb 2026 23:03:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Feb 2026 23:03:46 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Feb 2026 23:04:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 23:04:01 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 23:04:06 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 23:04:07 GMT
ENV GOLANG_VERSION=1.25.7
# Tue, 10 Feb 2026 23:05:32 GMT
RUN $url = 'https://dl.google.com/go/go1.25.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c75e5f4ff62d085cc0017be3ad19d5536f46825fa05db06ec468941f847e3228'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 23:05:33 GMT
WORKDIR C:\go
# Tue, 10 Feb 2026 23:32:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:32:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 10 Feb 2026 23:32:32 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 10 Feb 2026 23:32:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Feb 2026 23:32:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 10 Feb 2026 23:32:41 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf582aa59c8f589f6cc77378809eabf79b679ef8c09e8e900a5ce77bf0b77e38`  
		Last Modified: Tue, 10 Feb 2026 22:55:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6217e61f7864d34fd05bf54772d9c3b022ea829eae5ec0c5dab78956647dfdf`  
		Last Modified: Tue, 10 Feb 2026 23:05:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e899259ec619dc0a8102d6619bd89666cc46a2a3bbccc0b7c11d40b6a8f6754`  
		Last Modified: Tue, 10 Feb 2026 23:05:45 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb47edd4fee7b86824e8cc36311306f960e816acbca913485b6b9a80576e6b9`  
		Last Modified: Tue, 10 Feb 2026 23:05:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d98730645e41212165742bcb27dc3fd9c188f4748d1e1a99b368135f0ed59c`  
		Last Modified: Tue, 10 Feb 2026 23:05:44 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a0dd9893090f8a1293f5d2266ee7b61f09070fa1d0082dd3c138b9b9177205`  
		Last Modified: Tue, 10 Feb 2026 23:05:51 GMT  
		Size: 51.3 MB (51346334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7324a58e8872e7e77f36049b7e451f41fcbf8d404c35f0f03f6c70eee4434ab3`  
		Last Modified: Tue, 10 Feb 2026 23:05:43 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d86df17449bbcca695164e66e008ed5f7e61567528a81872e79544331682de`  
		Last Modified: Tue, 10 Feb 2026 23:05:43 GMT  
		Size: 339.2 KB (339164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c712947a99355861f1c83990bf00abd3e944cfe68bddeeeba881549c07f105`  
		Last Modified: Tue, 10 Feb 2026 23:05:43 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102a6ee71a8afce4a612a1eda8b9b8fea1f7bb40250371897f128420bd899e61`  
		Last Modified: Tue, 10 Feb 2026 23:05:54 GMT  
		Size: 62.6 MB (62570322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d43762dc4040c69eb5465d1aedee5985ec6a6c87d20c7f684aad08a6f342009`  
		Last Modified: Tue, 10 Feb 2026 23:05:43 GMT  
		Size: 1.5 KB (1460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b0951cdfa621025270840008d92efae57746b23e6999462027bf128935820`  
		Last Modified: Tue, 10 Feb 2026 23:32:46 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59cb7e1844f34da70c7880b91b4ac47dfa6ef68b408128df1fae65702f7f4e`  
		Last Modified: Tue, 10 Feb 2026 23:32:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d020d142a4e8fd36617f7ecb8c5c83df92e958851addb653373d7f37744e0a`  
		Last Modified: Tue, 10 Feb 2026 23:32:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce312b822bc5a3fe71c467373e8900bb6d67cb634061d9ef4a6bf643c237d50`  
		Last Modified: Tue, 10 Feb 2026 23:32:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86dcba59f1a290215a6b8f059ebe1931486a3950c21fa213901c473f27b8971`  
		Last Modified: Tue, 10 Feb 2026 23:32:45 GMT  
		Size: 2.3 MB (2291026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a665e187f4f465a4382ad9d49a05c312d1e64765f2193a88cbfdfd75716345`  
		Last Modified: Tue, 10 Feb 2026 23:32:45 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
