## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:86fb3f3b4ad13fc9e26300db1c539dcc0b1c33dfbfe31e9d6d6aacebcaaa8750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull caddy@sha256:2f6b4575eaaeb5a06d39a2c1129ca395e689ba1ac5e6995c794bcab2f9bf7fb5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2257123930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd3b32bbd01582ba5f453a455b631f987c68650612db6493707fef8a7568b7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:47:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:20 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Mar 2025 18:47:20 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Mar 2025 18:47:21 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Mar 2025 18:47:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Mar 2025 18:47:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:47:46 GMT
ENV GOPATH=C:\go
# Wed, 12 Mar 2025 18:47:53 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:47:53 GMT
ENV GOLANG_VERSION=1.23.7
# Wed, 12 Mar 2025 18:49:02 GMT
RUN $url = 'https://dl.google.com/go/go1.23.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'eba0477381037868738b47b0198d120a535eb9a8a17b2babb9ab0d5e912a2171'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:49:04 GMT
WORKDIR C:\go
# Wed, 12 Mar 2025 19:19:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:19:57 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 12 Mar 2025 19:19:58 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 12 Mar 2025 19:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 12 Mar 2025 19:20:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 12 Mar 2025 19:20:47 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca460218d31efd643af93062195cf5998927bbf927cec31d7b9cebba43204de0`  
		Last Modified: Wed, 12 Mar 2025 18:49:11 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe3d4affa0dda6481ab347a6ebb8e4459cc65ae99110a9a05ab7aa7447399e4`  
		Last Modified: Wed, 12 Mar 2025 18:49:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651cebcb94cdf1f075b6dba8df07bccdb2589c6e06fa2b7895242e28befd0843`  
		Last Modified: Wed, 12 Mar 2025 18:49:10 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240721af490884c9b2befc2789c6e5709c1145d52f310aa69535e5e4e74019ec`  
		Last Modified: Wed, 12 Mar 2025 18:49:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3012f7d8dada51682afbb93e6a336a0935cdb9cdab8789e1b03dfcad08561855`  
		Last Modified: Wed, 12 Mar 2025 18:49:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2265f412dc2a62819e66e26dd590b118fb6a0fb4aea77bbe9aea295e6151baa`  
		Last Modified: Wed, 12 Mar 2025 18:49:12 GMT  
		Size: 25.4 MB (25425495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91914f3905f9d2b849736011a0204df57019b199dfa24eb71d8485cbecdbaac3`  
		Last Modified: Wed, 12 Mar 2025 18:49:07 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97090ce4cd46329b41378283f83b2afc0437d223e3f407d7408cd8ed2686f9c5`  
		Last Modified: Wed, 12 Mar 2025 18:49:08 GMT  
		Size: 330.2 KB (330197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328093bcfae67a2fd2e71e460bfd855e02eac02db8c03d4ef4857644acc3f633`  
		Last Modified: Wed, 12 Mar 2025 18:49:07 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7ea6b2ecb26d2065939a2c659b413dcd295f8228623dfa864317c6160fb381`  
		Last Modified: Wed, 12 Mar 2025 18:49:19 GMT  
		Size: 77.4 MB (77427412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037d838db8570668af2cb061ae3f1ba62f39f002b21a86eec0fd3ab83dc396f2`  
		Last Modified: Wed, 12 Mar 2025 18:49:07 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad311ed7dcc05bf188631ee072e329d31ef541d125c55258c0891a617a5fe88e`  
		Last Modified: Wed, 12 Mar 2025 19:20:50 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c40ca941aff9a784c86f5588f376709466a562c560ccc9b2363172328d6f2`  
		Last Modified: Wed, 12 Mar 2025 19:20:49 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5694dff17587b9c868d39b28de8c4b3e93b731e31c72b5878ed072a85a6ad0`  
		Last Modified: Wed, 12 Mar 2025 19:20:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221058c9ca8eae4bf28849d8733df714e516c13a165ce0b762b53ca39a388a72`  
		Last Modified: Wed, 12 Mar 2025 19:20:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ad5f61b79dc10120a733e4782d8a4a828e6fea31402716114a5e374b04965e`  
		Last Modified: Wed, 12 Mar 2025 19:20:49 GMT  
		Size: 2.3 MB (2289132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a79935229be2be54b617bbc565dc20e5f2908f50eb17211b8b116a586f866f`  
		Last Modified: Wed, 12 Mar 2025 19:20:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
