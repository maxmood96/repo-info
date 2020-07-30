## `openjdk:8u265-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:89a6cd8e6d78333d4ed92beb41ded027cdf7696945a5275265f06de69ddfe107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:8u265-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:d99607ef0d6f5e17986545159aaf56eb6b0bdc519929898c5a2ed8a233429b26
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2424175150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c3f9f624cc905d60c9a0d01ce6e5dd772096c98d4520466663574d9dc3a0e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 02:27:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 29 Jul 2020 01:34:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 30 Jul 2020 22:15:58 GMT
ENV JAVA_VERSION=8u265
# Thu, 30 Jul 2020 22:15:59 GMT
ENV JAVA_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u265-b01/OpenJDK8U-jdk_x64_windows_8u265b01.zip
# Thu, 30 Jul 2020 22:17:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac -version'; javac -version; 	Write-Host '  java -version'; java -version; 		Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df9d9d4f1a50ee68e53390188a27d433831832a28f411a3139d70477d10675d`  
		Last Modified: Wed, 15 Jul 2020 02:53:31 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b3d7034be591a9d090e50c29e82c24fab7c18bfcca00ed67cdb92fa16b819e`  
		Last Modified: Wed, 29 Jul 2020 01:54:56 GMT  
		Size: 9.2 MB (9158120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e1a5c991cbf6c27388f85277556e3cd12c4994b2a3818ddd36a50ea98f5f39`  
		Last Modified: Thu, 30 Jul 2020 22:27:15 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9017a5345410bddbfaab10cb6c45fc1191d0c726fac526953a380f9fef689ed0`  
		Last Modified: Thu, 30 Jul 2020 22:27:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54831cfeaaa1224017afd33402f0d03d38616b237f20f169bf85c7fc1fee67d2`  
		Last Modified: Thu, 30 Jul 2020 22:27:29 GMT  
		Size: 104.8 MB (104820173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
