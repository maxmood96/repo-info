## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:f04e5383e566efe548c0546b5329a6046b1e2409c1fa097243d7de693aa49614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull caddy@sha256:715492b0f944cd127eb6bbb8a4c0cc689f7707fa7a5e2b472fc6452b4f07b90d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2398610240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c6d1145422423f4bf0e98d89ef4f0a046b691c5549c52870927143d9f07d39`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 07 Oct 2025 19:34:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 19:34:31 GMT
ENV GIT_VERSION=2.48.1
# Tue, 07 Oct 2025 19:34:33 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 07 Oct 2025 19:34:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 07 Oct 2025 19:34:35 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 07 Oct 2025 19:35:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:35:38 GMT
ENV GOPATH=C:\go
# Tue, 07 Oct 2025 19:35:44 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Oct 2025 19:35:44 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:37:16 GMT
RUN $url = 'https://dl.google.com/go/go1.25.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c18b46f6aa44dbfcd54a9db19dd2fcc5ad684819addcfcf968aa75dad89a89c8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:37:17 GMT
WORKDIR C:\go
# Tue, 07 Oct 2025 20:12:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 20:12:28 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Oct 2025 20:12:28 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 07 Oct 2025 20:12:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Oct 2025 20:12:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 Oct 2025 20:12:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84669fff65b3c9be81e40b9990f09af6d79236a36c89b48837a2c56193e23d4`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e60c3731686204945190028a490513225d391212a27fae945d09b2858d31e55`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d31081e3081cc502401b5490ba7207796e551806afd0270bd8a99cd079aeb`  
		Last Modified: Tue, 07 Oct 2025 19:46:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0ae39107ec10a072379114022d2a65f0876026a506d6d97879b0690375ff5a`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a9e7b99aa2b469a3ce0476da3574a6f1a3fd1a31ab60d087e3b241be8b602`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8795f0cd8577898069910151345b5cceb653b95293f0e07bd3ef305d4b319`  
		Last Modified: Tue, 07 Oct 2025 19:46:21 GMT  
		Size: 51.2 MB (51222673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b85e42e9abcbae149b2e2d9b074fa1b76e74cd88f54622eaef24b9ea51ab81`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d664c422bbdd3f488f9b864b914e4867001ad3abd4164492dce75542a29e954`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 353.6 KB (353616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3564e813d9de7e1f20fa71a8b4a152f09f76719c04ba40966f67fbefadab5d`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02b4977a05998859250a8498907467403796eda2afc717329e301fd821c6f1b`  
		Last Modified: Tue, 07 Oct 2025 19:46:41 GMT  
		Size: 62.6 MB (62575489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fb0b5a044068825be258eb2d74f38322a83d5679674bb7247d7c482011f670`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd774b4fe59f6b1be84c9ca72d0ec51480732efec0d929ef8e9b38c2a3fc89dc`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00883df518d9fb471f8a5583a0e58e0373a64e003dc5396513f3f766eec53d`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7881cce5aa1a5935de2405658071a0e5b1d9661b5487bc3c9aa9f53b6c5c10c1`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b38591ce3e10db96fe64de0a8ebc6f65514f302b2028d68b100a86fadde6d60`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aececf11534a88cf9a95165200a3a9f75ba72ec567775b4df9c7d596afc439f5`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 2.3 MB (2296303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efede2e44e94f6e665f2ecf900a0cd611dff2a029759937c9b5a480d4b3df131`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
