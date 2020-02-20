## `golang:windowsservercore`

```console
$ docker pull golang@sha256:e095e81f5e7e9ced4caea86fe84deff8f189bfc32dc09626bce64510030d4b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1040; amd64

### `golang:windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull golang@sha256:dd836044142e66a5478c413a3934208ba7c464412084de9ea5cb548ca31e998e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5902204818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ef4e4e8931568a1d11979029be98e189a1fa80c904cdf0eae4b812171c446d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 09:14:29 GMT
ENV GIT_VERSION=2.23.0
# Thu, 20 Feb 2020 09:14:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 20 Feb 2020 09:14:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 20 Feb 2020 09:14:33 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 20 Feb 2020 09:16:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 09:16:17 GMT
ENV GOPATH=C:\gopath
# Thu, 20 Feb 2020 09:17:39 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2020 09:38:17 GMT
ENV GOLANG_VERSION=1.13.8
# Thu, 20 Feb 2020 09:44:45 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'aaf0888907144ca7070c8dad03fcf1308f77a42d2f6e4d2a609e64e9ae73cf4f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 09:44:47 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560a5edc3b65548cd8f0a5736740259c10731b69be646647541d454f4a46d74d`  
		Last Modified: Thu, 20 Feb 2020 10:16:28 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d778cb1587245dbb3aa1eadff960d2ca6808181a7f76399e1461b4488dd0d110`  
		Last Modified: Thu, 20 Feb 2020 10:16:27 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc71d139522c2d69f799715a806ce8ce02bd536d9fb33c3c1cff0d512c06ebe`  
		Last Modified: Thu, 20 Feb 2020 10:16:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3aec6ae82f728acb67ab3203c9f84faf93c0ff671c1d1341837da6f6127ec3`  
		Last Modified: Thu, 20 Feb 2020 10:16:25 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6734e518b8f70059c148a428fbd47fe51d143e43477597a7b34afb502090a6cd`  
		Last Modified: Thu, 20 Feb 2020 10:16:57 GMT  
		Size: 30.5 MB (30460160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52c1cb26338697dbffd8fd282e956aa88db7f630a7b5c1c90f750eee04c24e4`  
		Last Modified: Thu, 20 Feb 2020 10:16:22 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58993efc965e34067a71381b74e269f61cff043dfd64a430cddfcd494cd3f21`  
		Last Modified: Thu, 20 Feb 2020 10:16:24 GMT  
		Size: 5.3 MB (5316014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1641e5e221d70fe47bdc6e53566f897cbacd924273c19d5103b8822eafb90b66`  
		Last Modified: Thu, 20 Feb 2020 10:23:23 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cab2aaa90d685cb58454410a4ce7a70ba56b5bce9527800358ab58e753bf66`  
		Last Modified: Thu, 20 Feb 2020 10:25:00 GMT  
		Size: 139.4 MB (139353947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a2c1a7c740886e212708af170a7b6a56680fd645dcde5257747f26f8454389`  
		Last Modified: Thu, 20 Feb 2020 10:23:22 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.17763.1040; amd64

```console
$ docker pull golang@sha256:712e12d23b76b9002033feac1ac078c8cf471ae40ab0ea77bfebacd9409cd6d6
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2390289417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24bb64f58e39afc52ee69b413bff6ed68fdac80cf04e44e4e30aecb99c38e21`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 09:24:51 GMT
ENV GIT_VERSION=2.23.0
# Thu, 20 Feb 2020 09:24:52 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 20 Feb 2020 09:24:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 20 Feb 2020 09:24:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 20 Feb 2020 09:26:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 09:26:04 GMT
ENV GOPATH=C:\gopath
# Thu, 20 Feb 2020 09:26:30 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 20 Feb 2020 09:45:07 GMT
ENV GOLANG_VERSION=1.13.8
# Thu, 20 Feb 2020 09:50:37 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'aaf0888907144ca7070c8dad03fcf1308f77a42d2f6e4d2a609e64e9ae73cf4f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 20 Feb 2020 09:50:39 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110dad01ccee3d09fea60ea0d52694e30fd66dde9aba2b80aecf974b583e715e`  
		Last Modified: Thu, 20 Feb 2020 10:18:49 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08227349fdb2e96c42cfe1dd8b9fc4d8a4a85e9a303fe293727eb01701bbcacf`  
		Last Modified: Thu, 20 Feb 2020 10:18:47 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fee65f96c94d8080d815d503bbc149109dd1f67641301deb251ab9473035e6`  
		Last Modified: Thu, 20 Feb 2020 10:18:47 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca5f0dbb9e1f23daefbfb48689ca6dbf034e885572be47a1ddab25dbd2daf2b`  
		Last Modified: Thu, 20 Feb 2020 10:18:47 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3010ef660c0462ec39174065b9aab710d1d830c63d271b91f0fa7ba9e7db38`  
		Last Modified: Thu, 20 Feb 2020 10:18:59 GMT  
		Size: 29.6 MB (29649597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1950846c735f1005e0ddd4a3bf964daa3d2b82a96afbbe1a9db1b1cfe95ad623`  
		Last Modified: Thu, 20 Feb 2020 10:18:44 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4aa2e260f5863265a5a10dd0bc9437eff66a067199e59f228354fa33138657`  
		Last Modified: Thu, 20 Feb 2020 10:18:44 GMT  
		Size: 294.9 KB (294889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17e46e643769eaf0144fdaa20baf3a135f6fb6e3221fa6b75746506fb0ead18`  
		Last Modified: Thu, 20 Feb 2020 10:25:44 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327a43cac0529e1998c0d4a992bfd9715e32a62e02681a3ffe9504989f602b29`  
		Last Modified: Thu, 20 Feb 2020 10:27:19 GMT  
		Size: 129.8 MB (129831322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44703b83db6fa112cd0af6796ab37546c1b70f54889c7290bc92fad2d94df98`  
		Last Modified: Thu, 20 Feb 2020 10:25:43 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
