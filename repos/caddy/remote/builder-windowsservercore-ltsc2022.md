## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:98d1fe44e4e2b37a766b9a036a3189825b88f9f2c5877ac67421adc54af0d088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull caddy@sha256:98e7acf808b1e43b79c8cb996dd188571ae45e8db4dde8729347621b3122edf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873763738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c381c2936d25a24d070de3ffd2ab13b3ee3ea8c09151213469404ddb673dcd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Jul 2023 20:29:19 GMT
ENV GIT_VERSION=2.23.0
# Thu, 13 Jul 2023 20:29:20 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 13 Jul 2023 20:29:21 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 13 Jul 2023 20:29:21 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 13 Jul 2023 20:30:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Jul 2023 20:30:03 GMT
ENV GOPATH=C:\go
# Thu, 13 Jul 2023 20:30:22 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Jul 2023 20:44:02 GMT
ENV GOLANG_VERSION=1.20.6
# Thu, 13 Jul 2023 20:46:22 GMT
RUN $url = 'https://dl.google.com/go/go1.20.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b67dd7f2b4589701e53c98e348e1b4d9a7c3536dc316941172b2f0b60ae4ce5f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Jul 2023 20:46:24 GMT
WORKDIR C:\go
# Fri, 14 Jul 2023 00:52:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:52:45 GMT
ENV XCADDY_VERSION=v0.3.4
# Mon, 17 Jul 2023 21:16:53 GMT
ENV CADDY_VERSION=v2.6.4
# Mon, 17 Jul 2023 21:16:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 17 Jul 2023 21:17:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('542b4c083852d41081186c79757b66ff3c26248f72ed461dbc038b51687d0a8a8ce8eee69e3b5a1d43360c48b3405b611b940fa378debe98aaa0b3c5aebfa218')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 17 Jul 2023 21:17:18 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ab322251f8c00d29baecc140e08d269c37b32475902e7a2822076226f616fa`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a968ab3b5ad50a23776f7dd7e039322644cac504ae091a0b0cd2e1b88fbb7e69`  
		Last Modified: Thu, 13 Jul 2023 21:07:34 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ba07cbbe0cde4ed464b5564160e204ded4877d3a1e5cf5fa3e155d5c0c3500`  
		Last Modified: Thu, 13 Jul 2023 21:07:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22efbf516ade60254b7399cfd7c01ac615e7d0c3745272b9636c39ba1b16c6e9`  
		Last Modified: Thu, 13 Jul 2023 21:07:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195ef065fa8b0419c3b6dc860031273f7cb1e3adab37c0a55458d916644f7f32`  
		Last Modified: Thu, 13 Jul 2023 21:07:40 GMT  
		Size: 25.5 MB (25535727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792bc8f98993f23c77f2a5ab339752f8bed1c5769eff7a72bd01f84cae18d978`  
		Last Modified: Thu, 13 Jul 2023 21:07:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ee2ce3d2ac713b0419f7347636dffe3f3d8639e4f3476fc6cf2f233ed3392b`  
		Last Modified: Thu, 13 Jul 2023 21:07:32 GMT  
		Size: 263.2 KB (263191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b68276445981c123966189306118e7fa72bbe151c38683372fa1818054c50c`  
		Last Modified: Thu, 13 Jul 2023 21:11:07 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635735e9f9d770e01c7a713c98765f3633e53c5280c4bccd2bda48b6a09af304`  
		Last Modified: Thu, 13 Jul 2023 21:11:30 GMT  
		Size: 108.9 MB (108905745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9299dfb70eb041a3dbae4b281918ddf3d544ade95ff70fdaae3b6fd6321c864c`  
		Last Modified: Thu, 13 Jul 2023 21:11:07 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4e73df4f4ff72ee78530a039696afe27847741d6825b02b348f360c5c58ded`  
		Last Modified: Fri, 14 Jul 2023 00:56:22 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa17ba2a6a63f370b02e694fdee8fafe232781cdf5a0541ba5d2bd563e140f6f`  
		Last Modified: Fri, 14 Jul 2023 00:56:20 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f062eb211d09374d403931f02beb6179dbc4ba6870d1bcf2c74b0a71b67d8c5`  
		Last Modified: Mon, 17 Jul 2023 21:23:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e307dd7f7673c44a3d3867b48076e6859d4a1883f3bf25cdeaa5e2f18d3639`  
		Last Modified: Mon, 17 Jul 2023 21:23:44 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1389e619134e9bc782f11430bda4dbd9ed60b4b012bf6f7efbc3682545905cd`  
		Last Modified: Mon, 17 Jul 2023 21:23:45 GMT  
		Size: 1.7 MB (1676101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664a0a46c98ef0d03ff2d96c35b1ab049acf1b7f43780628a41cd4801c63096c`  
		Last Modified: Mon, 17 Jul 2023 21:23:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
