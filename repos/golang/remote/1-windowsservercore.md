## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:71998d17ccbfd6bca172386203ae452f8617e7f422685cc647bceeb14a079641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `golang:1-windowsservercore` - windows version 10.0.26100.32995; amd64

```console
$ docker pull golang@sha256:8e89ed6ab1f1517e8d7c8622972f21d5178854e8577d95046853add89fcd4854
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2400723824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef9c399d83402d2aa12c65ec74a5d868464a1c3a9afc5ad5400b6453ec8c749`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:22:06 GMT
ENV GIT_VERSION=2.48.1
# Tue, 09 Jun 2026 22:22:06 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 09 Jun 2026 22:22:07 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 09 Jun 2026 22:22:08 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 09 Jun 2026 22:22:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:22:24 GMT
ENV GOPATH=C:\go
# Tue, 09 Jun 2026 22:22:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:22:31 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 09 Jun 2026 22:24:09 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:24:10 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde3f87c92fa7d0ae280c09db445ee43c8fe0d6469fc2c7ef39eccb597a279d6`  
		Last Modified: Tue, 09 Jun 2026 22:15:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272b25e4f9b588ef12b114aef37881b37bd4c18f895164f93fedb5b662d1214e`  
		Last Modified: Tue, 09 Jun 2026 22:24:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f95bbf2e19b06ae0fafacddcc2311a15a0e674639be5e9face2c87a623c5f6`  
		Last Modified: Tue, 09 Jun 2026 22:24:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd99af064001b3271c7db22a640bb6dd5ea71b5c34a6535fcae25a3502b626f9`  
		Last Modified: Tue, 09 Jun 2026 22:24:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb86163344ae33bad3e1f715047069c88dc758a5cb0b1bd7309d1be450f95b7`  
		Last Modified: Tue, 09 Jun 2026 22:24:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742b10c70845db0bb2dd0bf72ddb8a8c35425483635824b24bb3e380d7a676f5`  
		Last Modified: Tue, 09 Jun 2026 22:24:26 GMT  
		Size: 51.3 MB (51252538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5946af3e634fa1b8f9f213c3e22f7e86e4318880f7d7f9940df28595a9bf3b`  
		Last Modified: Tue, 09 Jun 2026 22:24:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dca8b428570c892454e9e7c960d09fec5e8cb4d7934dee10c4f27f229182c5`  
		Last Modified: Tue, 09 Jun 2026 22:24:19 GMT  
		Size: 383.5 KB (383489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456b6d42fed7962d0e86f03ef354a2e4c204796bdc66219dac933313cd2194dc`  
		Last Modified: Tue, 09 Jun 2026 22:24:18 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9db39ba4238180e591f9f214b990f235c8a6b6361066df530c7bd042bebd134`  
		Last Modified: Tue, 09 Jun 2026 22:24:30 GMT  
		Size: 69.9 MB (69934339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e77db804920b355a661f85c770aee26cd4a797c68ed868076d88e5533180ebe`  
		Last Modified: Tue, 09 Jun 2026 22:24:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull golang@sha256:e598fd6ad0f68efec0c4bd3b4d1ce7c3e595e49adde05b022d025499746e5b0a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2253721000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa676fc7991b4c54815146f48fd242670b51346b80a75d4f5cffe1d24904e540`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:21:21 GMT
ENV GIT_VERSION=2.48.1
# Tue, 09 Jun 2026 22:21:22 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 09 Jun 2026 22:21:22 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 09 Jun 2026 22:21:23 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 09 Jun 2026 22:21:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:21:44 GMT
ENV GOPATH=C:\go
# Tue, 09 Jun 2026 22:21:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:21:50 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 09 Jun 2026 22:23:21 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:23:22 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c9b713a469c080f684d10fd327070faf916b6d9b86f859442eebbd39bdd7b`  
		Last Modified: Tue, 09 Jun 2026 22:13:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a098369987f03c2a65b49ac10131cac211e11f761526867bcbe92d4b4dcd7b7`  
		Last Modified: Tue, 09 Jun 2026 22:23:29 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2fb521f36bd148a151bf309a42e68e1f8418888ca8decdf72f22d109ae1777`  
		Last Modified: Tue, 09 Jun 2026 22:23:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b4fd96a07dbe1a02824dfd2a4733cd9a665d217d2b392432605387bdc502df`  
		Last Modified: Tue, 09 Jun 2026 22:23:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84c8f6d0eb0eb93930aa98aa94c47965c17c041a9deffbfada31e22b25d8e6b`  
		Last Modified: Tue, 09 Jun 2026 22:23:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc51cb03e8ddded49624d9c63654845370ad0af9cebd295a8aa9d9ac25c8a55f`  
		Last Modified: Tue, 09 Jun 2026 22:23:34 GMT  
		Size: 51.3 MB (51344651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee856674db10ad35749acb48c1c240db61f308fb552766b57f0ba21a136b99`  
		Last Modified: Tue, 09 Jun 2026 22:23:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e04976cfb32755b87d94d48bb7b82955e1dd5c65f12905b83bb503d1935026`  
		Last Modified: Tue, 09 Jun 2026 22:23:26 GMT  
		Size: 339.5 KB (339467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6735a6f8b7e8ea333f742e2a89dddba3ccdc561ae45d2e93e65dfc3a31bae57`  
		Last Modified: Tue, 09 Jun 2026 22:23:26 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73bf2a8c2b226d10e07ee7391ca6365fd3ff721f9ecce769ad6d958119f7b07`  
		Last Modified: Tue, 09 Jun 2026 22:23:37 GMT  
		Size: 69.9 MB (69900705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c124c50e398aaa43b72fe40a5cc4950110b9196213c0c46b43973f1c418336`  
		Last Modified: Tue, 09 Jun 2026 22:23:26 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
