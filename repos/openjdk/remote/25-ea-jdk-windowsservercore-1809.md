## `openjdk:25-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:3ea058f1d1bd1dc16a7ad08213bf6e5eea75554d11515c7576f34bc15c05fbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:d9567d1e5a9d8b19acedfa085f2ce9f6e61b394746ae0e4dc475bcf4c6f2f631
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2223897539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b081d8d56dd1a009070589fbdab6155440fa65edc083e8628e28386d73d11456`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:41:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:42:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:41 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 11 Dec 2024 20:42:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:48 GMT
ENV JAVA_VERSION=25-ea+1
# Wed, 11 Dec 2024 20:42:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_windows-x64_bin.zip
# Wed, 11 Dec 2024 20:42:49 GMT
ENV JAVA_SHA256=e613057ce9dd454d410ac2462a504dd7679eeec29d28c18c9d16c6d12f12f346
# Wed, 11 Dec 2024 20:43:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:43:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3394029499f192ac3be229706271ea5e2d5a1604895ab66dab3173b9373fb981`  
		Last Modified: Wed, 11 Dec 2024 20:43:19 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b8d16b634861e5b13f96f4921e2c550ca0a7eb018c26ef965d81fa3603920e`  
		Last Modified: Wed, 11 Dec 2024 20:43:19 GMT  
		Size: 473.2 KB (473233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d836079c7592f6d11730f7646bc82fe68ada389debefc31808e74b7f9d5077`  
		Last Modified: Wed, 11 Dec 2024 20:43:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae3ef5e1a6e39e83daae8ab302782353f59ea0f7cf3a8c247522ca7ee4f90a3`  
		Last Modified: Wed, 11 Dec 2024 20:43:19 GMT  
		Size: 324.3 KB (324277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9c106f4166a57968bb01c1d3ef094f968de477b1c7b228101eb2784726d00c`  
		Last Modified: Wed, 11 Dec 2024 20:43:18 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7830650946fc8d807cd0994465d345837d22a10fa0f231c07efaf0a1e3686e`  
		Last Modified: Wed, 11 Dec 2024 20:43:18 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808f35b3c5234c6275017242c38c8fbcb3477ca1978eaecd5aa0de0ee1d10faa`  
		Last Modified: Wed, 11 Dec 2024 20:43:18 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8073c63f315cb2646f01cdb3afdd37a8a8eaedad39645062476c68a90b50bde4`  
		Last Modified: Wed, 11 Dec 2024 20:43:30 GMT  
		Size: 208.9 MB (208922057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f59074833366a6d0cb0b81fbe5de0eae346f9b68bf6cb263bb855386b3439bc`  
		Last Modified: Wed, 11 Dec 2024 20:43:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
