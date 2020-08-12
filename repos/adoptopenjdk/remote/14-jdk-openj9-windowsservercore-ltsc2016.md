## `adoptopenjdk:14-jdk-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:72a0e09dbf2703458bad507c2eda83bb6c609f90b0ef18bb794ad54a71f234af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `adoptopenjdk:14-jdk-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull adoptopenjdk@sha256:3106c614ea251794d3bf0ef204e8c77e468fa3cb3f94d1c09595748db67884fa
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6132447285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321b4da12d73868b3e159030212cd46521f2c2152b3236d3226c3741eaf4b8c3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 17:34:23 GMT
ENV JAVA_VERSION=jdk-14.0.2+12_openj9-0.21.0
# Wed, 12 Aug 2020 17:37:34 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12_openj9-0.21.0/OpenJDK14U-jdk_x64_windows_openj9_14.0.2_12_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12_openj9-0.21.0/OpenJDK14U-jdk_x64_windows_openj9_14.0.2_12_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (2e496ce7ca02f7a380fd1902e06d55d52121bb2eee29b21b8e54ad3e2fd3466e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2e496ce7ca02f7a380fd1902e06d55d52121bb2eee29b21b8e54ad3e2fd3466e') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 17:37:35 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 12 Aug 2020 17:37:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789d769583cce17c20c6237588a7064b7069fd8429f787e852100daeb0ebd9f`  
		Last Modified: Wed, 12 Aug 2020 18:13:14 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1a15bff823e4f7f79790a0d2d174179d64a0c2c445b53fa6383813039e2301`  
		Last Modified: Wed, 12 Aug 2020 18:14:11 GMT  
		Size: 394.3 MB (394295241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31967ee0d8c232da1e1c6ef748f180e3f9b693a0a2be2d6063a02fdda95bc11f`  
		Last Modified: Wed, 12 Aug 2020 18:13:14 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a704eb8b811eae9844e1a0744b9d45f9f2987404cb17fe0c351f717a1eaaf6af`  
		Last Modified: Wed, 12 Aug 2020 18:13:14 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
