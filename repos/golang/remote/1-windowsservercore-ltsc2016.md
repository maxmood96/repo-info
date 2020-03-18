## `golang:1-windowsservercore-ltsc2016`

```console
$ docker pull golang@sha256:e6096bb03e64a2cef46ff8e98fa02170ff6cf2d04230162bb6bf2596f7cb05fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `golang:1-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull golang@sha256:b52dfa750ab6143744f4a33ef2eade06ee8919e07feccb8edff0c97a2fbbe010
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5907372892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9d8f691f10027f37fce137c2078fa935991a9c75af9881e62f99b0f3095385`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Mar 2020 12:12:50 GMT
ENV GIT_VERSION=2.23.0
# Wed, 18 Mar 2020 12:12:51 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 18 Mar 2020 12:12:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 18 Mar 2020 12:12:53 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 18 Mar 2020 12:14:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 18 Mar 2020 12:14:16 GMT
ENV GOPATH=C:\gopath
# Wed, 18 Mar 2020 12:15:28 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 18 Mar 2020 12:15:29 GMT
ENV GOLANG_VERSION=1.14
# Wed, 18 Mar 2020 12:19:06 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cc2f1e8d19744fe0b2e979bf9a4f9d224e416f4f54cb6cf3aa8b5e9c0865de37'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 18 Mar 2020 12:19:08 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f08cc5bf7287bc1d8f72edfe2439c99210e433230a22fc73264fcf1685850ed2`  
		Last Modified: Fri, 13 Mar 2020 22:09:47 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d561174ac001ca0d7adb9545849bd36e269ed33f40531a998720c250c43ffb`  
		Last Modified: Wed, 18 Mar 2020 12:23:55 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d21a03a688a549f1ddaa9d9d5bb998cb8a2c0e9788b802541787ca3f1ed8ff8`  
		Last Modified: Wed, 18 Mar 2020 12:23:53 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4d91f9428f64df474729562c61ed53946510b7ab35a33f254d5cae955259ba`  
		Last Modified: Wed, 18 Mar 2020 12:23:52 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd05a2f1cca3f7d532ddb895f160f78d4de3724c6ffcf07015232115e4a95f`  
		Last Modified: Wed, 18 Mar 2020 12:23:52 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8427dcc64be825a40aa719b7fa0062a8c227563d3d6e47a4239ea5e013d65401`  
		Last Modified: Wed, 18 Mar 2020 12:23:57 GMT  
		Size: 30.5 MB (30489302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45815090f3ebeaafd58a49c3138251d3bccaaa64ff19dfdf4e7f9c3ac65fd10`  
		Last Modified: Wed, 18 Mar 2020 12:23:49 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009d25c2b0e7b36367e585fa0ea36993bf6e78051273a0e15e8251aff32436ad`  
		Last Modified: Wed, 18 Mar 2020 12:23:50 GMT  
		Size: 5.4 MB (5379505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce565c4e46ed83e9949538111c3ba2e4f4fc83ab5f0f696a20f59275d3c21fb2`  
		Last Modified: Wed, 18 Mar 2020 12:23:49 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e01cc3be0cf7da4338c54b1f62ac80a53bdb42d161bbf6985b7dad1adf58c`  
		Last Modified: Wed, 18 Mar 2020 12:26:09 GMT  
		Size: 142.7 MB (142733797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed431d009ee8fe6c0a15b776207ee5bd8d823ae364dbb63814f2b84e189266a`  
		Last Modified: Wed, 18 Mar 2020 12:23:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
